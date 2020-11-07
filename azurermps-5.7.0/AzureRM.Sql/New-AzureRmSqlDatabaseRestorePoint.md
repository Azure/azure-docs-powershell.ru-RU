---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseRestorePoint.md
ms.openlocfilehash: 1305e9e74b0f8a2ef1a8d866d4a2dd6d62e1cef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733537"
---
# <span data-ttu-id="ae3cb-101">New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ae3cb-101">New-AzureRmSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="ae3cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae3cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3cb-103">Создает новую точку восстановления, из которой можно восстановить базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae3cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae3cb-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae3cb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae3cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ae3cb-106">Командлет **New-AzureRmSqlDatabaseRestorePoint** создает новую точку восстановления, из которой можно восстановить базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-106">The **New-AzureRmSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Database can be restored from.</span></span>

<span data-ttu-id="ae3cb-107">Этот командлет в настоящее время поддерживается службой хранилища данных SQL Server в Azure.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-107">This cmdlet is currently supported by the SQL Server Datawarehouse service on Azure SQL Database.</span></span>

## <span data-ttu-id="ae3cb-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae3cb-108">EXAMPLES</span></span>

### <span data-ttu-id="ae3cb-109">Пример 1: создание точки восстановления</span><span class="sxs-lookup"><span data-stu-id="ae3cb-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzureRmSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="ae3cb-110">Эта команда создает точку восстановления для базы данных SQL Azure и возвращает сведения о точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-110">This command creates a restore point for Azure SQL Database and returns the details of the restore point.</span></span>

## <span data-ttu-id="ae3cb-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae3cb-111">PARAMETERS</span></span>

### <span data-ttu-id="ae3cb-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae3cb-112">-DatabaseName</span></span>
<span data-ttu-id="ae3cb-113">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="ae3cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3cb-114">-DefaultProfile</span></span>
<span data-ttu-id="ae3cb-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ae3cb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae3cb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae3cb-116">-ResourceGroupName</span></span>
<span data-ttu-id="ae3cb-117">Указывает имя группы ресурсов, которой назначена база данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="ae3cb-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="ae3cb-118">-RestorePointLabel</span></span>
<span data-ttu-id="ae3cb-119">Задает метку точки восстановления для упрощения идентификации.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae3cb-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ae3cb-120">-ServerName</span></span>
<span data-ttu-id="ae3cb-121">Указывает имя сервера AzureSQL, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="ae3cb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae3cb-122">-Confirm</span></span>
<span data-ttu-id="ae3cb-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae3cb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae3cb-124">-WhatIf</span></span>
<span data-ttu-id="ae3cb-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae3cb-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae3cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3cb-127">CommonParameters</span></span>
<span data-ttu-id="ae3cb-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae3cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3cb-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae3cb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3cb-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae3cb-130">INPUTS</span></span>

## <span data-ttu-id="ae3cb-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae3cb-131">OUTPUTS</span></span>

## <span data-ttu-id="ae3cb-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae3cb-132">NOTES</span></span>

## <span data-ttu-id="ae3cb-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae3cb-133">RELATED LINKS</span></span>
