---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1C0AF5B2-7187-4BFA-8DBB-A771FD2E00A4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: a4538210c95f8357a9b920f827e8812b47377a2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562056"
---
# <span data-ttu-id="2cd12-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2cd12-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="2cd12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cd12-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd12-103">Возвращает политику хранения для базы данных с долговременным сохранением.</span><span class="sxs-lookup"><span data-stu-id="2cd12-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cd12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cd12-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cd12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cd12-105">DESCRIPTION</span></span>
<span data-ttu-id="2cd12-106">Командлет **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** получает долгосрочную политику хранения, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="2cd12-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="2cd12-107">Политика — это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="2cd12-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="2cd12-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cd12-108">EXAMPLES</span></span>

## <span data-ttu-id="2cd12-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cd12-109">PARAMETERS</span></span>

### <span data-ttu-id="2cd12-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2cd12-110">-DatabaseName</span></span>
<span data-ttu-id="2cd12-111">Указывает имя базы данных SQL, для которой этот командлет получает политику.</span><span class="sxs-lookup"><span data-stu-id="2cd12-111">Specifies the name of the SQL Database for which this cmdlet gets a policy.</span></span>

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

### <span data-ttu-id="2cd12-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd12-112">-ResourceGroupName</span></span>
<span data-ttu-id="2cd12-113">Указывает имя группы ресурсов, содержащей базу данных.</span><span class="sxs-lookup"><span data-stu-id="2cd12-113">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="2cd12-114">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2cd12-114">-ServerName</span></span>
<span data-ttu-id="2cd12-115">Указывает сервер, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="2cd12-115">Specifies the server that hosts the database.</span></span>

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

### <span data-ttu-id="2cd12-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cd12-116">-Confirm</span></span>
<span data-ttu-id="2cd12-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2cd12-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cd12-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cd12-118">-WhatIf</span></span>
<span data-ttu-id="2cd12-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2cd12-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cd12-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2cd12-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cd12-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd12-121">-DefaultProfile</span></span>
<span data-ttu-id="2cd12-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cd12-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cd12-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd12-123">CommonParameters</span></span>
<span data-ttu-id="2cd12-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cd12-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd12-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cd12-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd12-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cd12-126">INPUTS</span></span>

## <span data-ttu-id="2cd12-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cd12-127">OUTPUTS</span></span>

## <span data-ttu-id="2cd12-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cd12-128">NOTES</span></span>

## <span data-ttu-id="2cd12-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cd12-129">RELATED LINKS</span></span>

[<span data-ttu-id="2cd12-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2cd12-130">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2cd12-131">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2cd12-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
