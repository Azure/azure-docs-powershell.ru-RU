---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: cb3cf5ee27afff0f95d1d649ec955a136cb76dba
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419292"
---
# <span data-ttu-id="3047f-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="3047f-101">Get-AzSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="3047f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3047f-102">SYNOPSIS</span></span>
<span data-ttu-id="3047f-103">Возвращает ход сканирования базы данных по TDE.</span><span class="sxs-lookup"><span data-stu-id="3047f-103">Gets the progress of a TDE scan of a database.</span></span>

## <span data-ttu-id="3047f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3047f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3047f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3047f-105">DESCRIPTION</span></span>
<span data-ttu-id="3047f-106">Для выполнения проверки прозрачного шифрования данных (TDE) в базе данных Azure SQL используется **cmdlet Get-AzSqlDataTransparentDataEncryptionActivity.**</span><span class="sxs-lookup"><span data-stu-id="3047f-106">The **Get-AzSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="3047f-107">Если диапазон шифрования не используется, этот cmdlet возвращает пустой список.</span><span class="sxs-lookup"><span data-stu-id="3047f-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="3047f-108">Дополнительные сведения см. в теме "Прозрачное шифрование данных с помощью SQL Azure "База данных" https://msdn.microsoft.com/library/dn948096 https://msdn.microsoft.com/library/dn948096) (Microsoft Developer Network библиотеки).</span><span class="sxs-lookup"><span data-stu-id="3047f-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>
<span data-ttu-id="3047f-109">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="3047f-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3047f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3047f-110">EXAMPLES</span></span>

### <span data-ttu-id="3047f-111">Пример 1. Получить действие TDE для базы данных</span><span class="sxs-lookup"><span data-stu-id="3047f-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="3047f-112">Эта команда возвращает действие TDE для базы данных database01 на сервере с именем server01.</span><span class="sxs-lookup"><span data-stu-id="3047f-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="3047f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3047f-113">PARAMETERS</span></span>

### <span data-ttu-id="3047f-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3047f-114">-DatabaseName</span></span>
<span data-ttu-id="3047f-115">Имя базы данных, для которой этот cmdlet получает шифрование TDE.</span><span class="sxs-lookup"><span data-stu-id="3047f-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="3047f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3047f-116">-DefaultProfile</span></span>
<span data-ttu-id="3047f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3047f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3047f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3047f-118">-ResourceGroupName</span></span>
<span data-ttu-id="3047f-119">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="3047f-119">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="3047f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3047f-120">-ServerName</span></span>
<span data-ttu-id="3047f-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3047f-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="3047f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3047f-122">-Confirm</span></span>
<span data-ttu-id="3047f-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3047f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3047f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3047f-124">-WhatIf</span></span>
<span data-ttu-id="3047f-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3047f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3047f-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3047f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3047f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3047f-127">CommonParameters</span></span>
<span data-ttu-id="3047f-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3047f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3047f-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3047f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3047f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3047f-130">INPUTS</span></span>

### <span data-ttu-id="3047f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3047f-131">System.String</span></span>

## <span data-ttu-id="3047f-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3047f-132">OUTPUTS</span></span>

### <span data-ttu-id="3047f-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="3047f-133">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="3047f-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3047f-134">NOTES</span></span>

## <span data-ttu-id="3047f-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3047f-135">RELATED LINKS</span></span>

[<span data-ttu-id="3047f-136">Get-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3047f-136">Get-AzSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="3047f-137">Set-AzSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="3047f-137">Set-AzSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzSqlDatabaseTransparentDataEncryption.md)


