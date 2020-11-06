---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2328631F-BC30-40E3-ADF7-B1D3B46A6E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryption.md
ms.openlocfilehash: 0566396e3a32891b010b2bfa3cd71ba47d4a7e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560427"
---
# <span data-ttu-id="9f401-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="9f401-101">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>

## <span data-ttu-id="9f401-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f401-102">SYNOPSIS</span></span>
<span data-ttu-id="9f401-103">Возвращает состояние TDE для базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f401-103">Gets the TDE state for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f401-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f401-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryption [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9f401-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f401-105">DESCRIPTION</span></span>
<span data-ttu-id="9f401-106">Командлет **Get-AzureRmSqlDatabaseTransparentDataEncryption** получает состояние прозрачного шифрования данных (TDE) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9f401-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure SQL database.</span></span>
<span data-ttu-id="9f401-107">Дополнительные сведения можно найти в разделе прозрачное шифрование данных с базой данных Azure SQL https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) в сетевой библиотеке разработчиков Microsoft).</span><span class="sxs-lookup"><span data-stu-id="9f401-107">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="9f401-108">Этот командлет получает текущее состояние TDE, но как шифрование, так и расшифровка могут быть долго выполняющимися операциями.</span><span class="sxs-lookup"><span data-stu-id="9f401-108">This cmdlet gets the current state of TDE, but both encryption and decryption can be long-running operations.</span></span>
<span data-ttu-id="9f401-109">Чтобы просмотреть процесс проверки шифрования, запустите командлет Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.</span><span class="sxs-lookup"><span data-stu-id="9f401-109">To see the encryption scan progress, run the Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity cmdlet.</span></span>

<span data-ttu-id="9f401-110">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="9f401-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9f401-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f401-111">EXAMPLES</span></span>

### <span data-ttu-id="9f401-112">Пример 1: получение состояния TDE для базы данных</span><span class="sxs-lookup"><span data-stu-id="9f401-112">Example 1: Get TDE status for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryption -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName             ServerName                    DatabaseName                                          State
-----------------             ----------                    ------------                                          -----
resourcegroup01               server01                      database01                                            Disabled
```

<span data-ttu-id="9f401-113">Эта команда получает состояние TDE для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="9f401-113">This command gets the status of TDE for the database named Database01 on the server named server01.</span></span>

## <span data-ttu-id="9f401-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f401-114">PARAMETERS</span></span>

### <span data-ttu-id="9f401-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9f401-115">-DatabaseName</span></span>
<span data-ttu-id="9f401-116">Указывает имя базы данных, для которой этот командлет получает состояние TDE.</span><span class="sxs-lookup"><span data-stu-id="9f401-116">Specifies the name of the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="9f401-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f401-117">-ResourceGroupName</span></span>
<span data-ttu-id="9f401-118">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="9f401-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9f401-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9f401-119">-ServerName</span></span>
<span data-ttu-id="9f401-120">Указывает имя сервера, на котором размещается база данных, для которой этот командлет получает состояние TDE.</span><span class="sxs-lookup"><span data-stu-id="9f401-120">Specifies the name of the server that hosts the database for which this cmdlet gets TDE status.</span></span>

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

### <span data-ttu-id="9f401-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f401-121">-Confirm</span></span>
<span data-ttu-id="9f401-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f401-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f401-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f401-123">-WhatIf</span></span>
<span data-ttu-id="9f401-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f401-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f401-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f401-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f401-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f401-126">-DefaultProfile</span></span>
<span data-ttu-id="9f401-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f401-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f401-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f401-128">CommonParameters</span></span>
<span data-ttu-id="9f401-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f401-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f401-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f401-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f401-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f401-131">INPUTS</span></span>

## <span data-ttu-id="9f401-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f401-132">OUTPUTS</span></span>

### <span data-ttu-id="9f401-133">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionModel</span><span class="sxs-lookup"><span data-stu-id="9f401-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionModel</span></span>

## <span data-ttu-id="9f401-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f401-134">NOTES</span></span>

## <span data-ttu-id="9f401-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f401-135">RELATED LINKS</span></span>

[<span data-ttu-id="9f401-136">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="9f401-136">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md)

[<span data-ttu-id="9f401-137">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="9f401-137">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)
