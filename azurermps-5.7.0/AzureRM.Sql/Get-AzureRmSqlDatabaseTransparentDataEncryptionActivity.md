---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7506FCEC-F96C-4918-8F20-A4B260F4DE1C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasetransparentdataencryptionactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity.md
ms.openlocfilehash: ec7c452939d82b82deed507c667bdc9cdeab3cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566084"
---
# <span data-ttu-id="dd1b6-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span><span class="sxs-lookup"><span data-stu-id="dd1b6-101">Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity</span></span>

## <span data-ttu-id="dd1b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd1b6-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1b6-103">Получает ход выполнения сканирования TDE базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-103">Gets the progress of a TDE scan of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd1b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd1b6-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd1b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd1b6-105">DESCRIPTION</span></span>
<span data-ttu-id="dd1b6-106">Командлет **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** получает сведения о ходе выполнения проверки прозрачного шифрования данных (TDE) для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-106">The **Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity** cmdlet gets the progress of a Transparent Data Encryption (TDE) scan of an Azure SQL database.</span></span>
<span data-ttu-id="dd1b6-107">Если диапазон шифрования не выполняется, этот командлет возвращает пустой список.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-107">If no encryption span is running, this cmdlet returns an empty list.</span></span>
<span data-ttu-id="dd1b6-108">Дополнительные сведения можно найти в разделе прозрачное шифрование данных с базой данных Azure SQL https://msdn.microsoft.com/library/dn948096 ( https://msdn.microsoft.com/library/dn948096) в сетевой библиотеке разработчиков Microsoft).</span><span class="sxs-lookup"><span data-stu-id="dd1b6-108">For more information, see Transparent Data Encryption with Azure SQL Databasehttps://msdn.microsoft.com/library/dn948096 (https://msdn.microsoft.com/library/dn948096) in the Microsoft Developer Network Library.</span></span>

<span data-ttu-id="dd1b6-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="dd1b6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd1b6-110">EXAMPLES</span></span>

### <span data-ttu-id="dd1b6-111">Пример 1: получение TDE действия для базы данных</span><span class="sxs-lookup"><span data-stu-id="dd1b6-111">Example 1: Get TDE activity for a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseTransparentDataEncryptionActivity -ServerName "server01" -ResourceGroupName "resourcegroup01" -DatabaseName "database01"
ResourceGroupName : resourcegroup01
ServerName        : server01
DatabaseName      : database01
Status            : Encrypting
PercentComplete   : 3.662109
```

<span data-ttu-id="dd1b6-112">Эта команда получает действие TDE для базы данных с именем Database01 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-112">This command gets the TDE activity for the database named database01 on the server named server01.</span></span>

## <span data-ttu-id="dd1b6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd1b6-113">PARAMETERS</span></span>

### <span data-ttu-id="dd1b6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd1b6-114">-DatabaseName</span></span>
<span data-ttu-id="dd1b6-115">Указывает имя базы данных, для которой этот командлет получает TDE шифрование.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-115">Specifies the name of the database for which this cmdlet gets TDE encryption activity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1b6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1b6-116">-DefaultProfile</span></span>
<span data-ttu-id="dd1b6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd1b6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd1b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd1b6-119">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-119">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1b6-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="dd1b6-120">-ServerName</span></span>
<span data-ttu-id="dd1b6-121">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-121">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1b6-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd1b6-122">-Confirm</span></span>
<span data-ttu-id="dd1b6-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1b6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd1b6-124">-WhatIf</span></span>
<span data-ttu-id="dd1b6-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd1b6-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd1b6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1b6-127">CommonParameters</span></span>
<span data-ttu-id="dd1b6-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1b6-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd1b6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1b6-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd1b6-130">INPUTS</span></span>

### <span data-ttu-id="dd1b6-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="dd1b6-131">None</span></span>
<span data-ttu-id="dd1b6-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="dd1b6-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dd1b6-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd1b6-133">OUTPUTS</span></span>

### <span data-ttu-id="dd1b6-134">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureSqlDatabaseTransparentDataEncryptionActivityModel</span><span class="sxs-lookup"><span data-stu-id="dd1b6-134">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlDatabaseTransparentDataEncryptionActivityModel</span></span>

## <span data-ttu-id="dd1b6-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd1b6-135">NOTES</span></span>

## <span data-ttu-id="dd1b6-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd1b6-136">RELATED LINKS</span></span>

[<span data-ttu-id="dd1b6-137">Get-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="dd1b6-137">Get-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Get-AzureRmSqlDatabaseTransparentDataEncryption.md)

[<span data-ttu-id="dd1b6-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="dd1b6-138">Set-AzureRmSqlDatabaseTransparentDataEncryption</span></span>](./Set-AzureRmSqlDatabaseTransparentDataEncryption.md)


