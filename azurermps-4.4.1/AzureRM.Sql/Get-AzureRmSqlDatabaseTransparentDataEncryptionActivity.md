---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: 0f858e2ad0260995b71ec6146a6ce7e64bd48c29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732269"
---
# <span data-ttu-id="4e4a8-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="4e4a8-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="4e4a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e4a8-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4a8-103">Получает ход выполнения сканирования TDE базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e4a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e4a8-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e4a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e4a8-105">DESCRIPTION</span></span>
<span data-ttu-id="4e4a8-106">Командлет **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** получает сведения о ходе выполнения проверки прозрачного шифрования данных (TDE) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="4e4a8-107">Если диапазон шифрования не выполняется, этот командлет возвращает пустой список.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="4e4a8-108">Дополнительные сведения можно найти в разделе прозрачное шифрование данных с базой данных Azure SQL https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) в сетевой библиотеке разработчиков Microsoft).</span><span class="sxs-lookup"><span data-stu-id="4e4a8-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="4e4a8-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4e4a8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e4a8-110">EXAMPLES</span></span>

### <span data-ttu-id="4e4a8-111">Пример 1: получение TDE действия для базы данных</span><span class="sxs-lookup"><span data-stu-id="4e4a8-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="4e4a8-112">Эта команда получает действие TDE для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="4e4a8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e4a8-113">PARAMETERS</span></span>

### <span data-ttu-id="4e4a8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e4a8-114">-DatabaseName</span></span>
<span data-ttu-id="4e4a8-115">Указывает имя базы данных, для которой этот командлет получает TDE шифрование.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

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

### <span data-ttu-id="4e4a8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e4a8-116">-ResourceGroupName</span></span>
<span data-ttu-id="4e4a8-117">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-117">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4e4a8-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4e4a8-118">-ServerName</span></span>
<span data-ttu-id="4e4a8-119">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="4e4a8-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e4a8-120">-Confirm</span></span>
<span data-ttu-id="4e4a8-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e4a8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4a8-122">-WhatIf</span></span>
<span data-ttu-id="4e4a8-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4a8-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e4a8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4a8-125">-DefaultProfile</span></span>
<span data-ttu-id="4e4a8-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e4a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4a8-127">CommonParameters</span></span>
<span data-ttu-id="4e4a8-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e4a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4a8-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e4a8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4a8-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e4a8-130">INPUTS</span></span>

## <span data-ttu-id="4e4a8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e4a8-131">OUTPUTS</span></span>

### <span data-ttu-id="4e4a8-132">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="4e4a8-132">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="4e4a8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e4a8-133">NOTES</span></span>

## <span data-ttu-id="4e4a8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e4a8-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e4a8-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4e4a8-135">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="4e4a8-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4e4a8-136">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


