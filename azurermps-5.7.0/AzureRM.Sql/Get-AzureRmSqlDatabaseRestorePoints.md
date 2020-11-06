---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaserestorepoints
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: fac0e279bb52ecf17246926875daea4392e23e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566091"
---
# <span data-ttu-id="82b9a-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="82b9a-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="82b9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82b9a-102">SYNOPSIS</span></span>
<span data-ttu-id="82b9a-103">Извлекает различные точки восстановления, из которых может быть восстановлено хранилище данных SQL.</span><span class="sxs-lookup"><span data-stu-id="82b9a-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82b9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82b9a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82b9a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b9a-105">DESCRIPTION</span></span>
<span data-ttu-id="82b9a-106">Командлет **Get-AzureRmSqlDatabaseRestorePoints** извлекает отдельные точки восстановления, из которых может быть восстановлено хранилище данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="82b9a-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="82b9a-107">Для базы данных SQL Azure окно восстановления непрерывно.</span><span class="sxs-lookup"><span data-stu-id="82b9a-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="82b9a-108">Это означает, что в качестве точки восстановления можно использовать любой момент времени в течение срока хранения резервной копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="82b9a-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>

<span data-ttu-id="82b9a-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="82b9a-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="82b9a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82b9a-110">EXAMPLES</span></span>

### <span data-ttu-id="82b9a-111">Пример 1: получение всех точек восстановления</span><span class="sxs-lookup"><span data-stu-id="82b9a-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="82b9a-112">Эта команда возвращает все доступные точки восстановления для базы данных SQL Azure с именем Database01.</span><span class="sxs-lookup"><span data-stu-id="82b9a-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="82b9a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82b9a-113">PARAMETERS</span></span>

### <span data-ttu-id="82b9a-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="82b9a-114">-DatabaseName</span></span>
<span data-ttu-id="82b9a-115">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="82b9a-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="82b9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b9a-116">-DefaultProfile</span></span>
<span data-ttu-id="82b9a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82b9a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82b9a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b9a-118">-ResourceGroupName</span></span>
<span data-ttu-id="82b9a-119">Указывает имя группы ресурсов, которой назначена база данных SQL.</span><span class="sxs-lookup"><span data-stu-id="82b9a-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="82b9a-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="82b9a-120">-ServerName</span></span>
<span data-ttu-id="82b9a-121">Указывает имя сервера AzureSQL, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="82b9a-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="82b9a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82b9a-122">-Confirm</span></span>
<span data-ttu-id="82b9a-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="82b9a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82b9a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82b9a-124">-WhatIf</span></span>
<span data-ttu-id="82b9a-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="82b9a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82b9a-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="82b9a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82b9a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b9a-127">CommonParameters</span></span>
<span data-ttu-id="82b9a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82b9a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b9a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82b9a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b9a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82b9a-130">INPUTS</span></span>

### <span data-ttu-id="82b9a-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="82b9a-131">None</span></span>
<span data-ttu-id="82b9a-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="82b9a-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82b9a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82b9a-133">OUTPUTS</span></span>

## <span data-ttu-id="82b9a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="82b9a-134">NOTES</span></span>

## <span data-ttu-id="82b9a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82b9a-135">RELATED LINKS</span></span>
