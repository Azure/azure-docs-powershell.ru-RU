---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseRestorePoints.md
ms.openlocfilehash: 002b248195840cb7453757e92f9269e7a61d9fda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566268"
---
# <span data-ttu-id="ffba9-101">Get-AzureRmSqlDatabaseRestorePoints</span><span class="sxs-lookup"><span data-stu-id="ffba9-101">Get-AzureRmSqlDatabaseRestorePoints</span></span>

## <span data-ttu-id="ffba9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffba9-102">SYNOPSIS</span></span>
<span data-ttu-id="ffba9-103">Извлекает различные точки восстановления, из которых может быть восстановлено хранилище данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ffba9-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffba9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffba9-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseRestorePoints [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffba9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffba9-105">DESCRIPTION</span></span>
<span data-ttu-id="ffba9-106">Командлет **Get-AzureRmSqlDatabaseRestorePoints** извлекает отдельные точки восстановления, из которых может быть восстановлено хранилище данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ffba9-106">The **Get-AzureRmSqlDatabaseRestorePoints** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="ffba9-107">Для базы данных SQL Azure окно восстановления непрерывно.</span><span class="sxs-lookup"><span data-stu-id="ffba9-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="ffba9-108">Это означает, что в качестве точки восстановления можно использовать любой момент времени в течение срока хранения резервной копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="ffba9-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>

<span data-ttu-id="ffba9-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="ffba9-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ffba9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffba9-110">EXAMPLES</span></span>

### <span data-ttu-id="ffba9-111">Пример 1: получение всех точек восстановления</span><span class="sxs-lookup"><span data-stu-id="ffba9-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseRestorePoints -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
```

<span data-ttu-id="ffba9-112">Эта команда возвращает все доступные точки восстановления для базы данных SQL Azure с именем Database01.</span><span class="sxs-lookup"><span data-stu-id="ffba9-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="ffba9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffba9-113">PARAMETERS</span></span>

### <span data-ttu-id="ffba9-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ffba9-114">-DatabaseName</span></span>
<span data-ttu-id="ffba9-115">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ffba9-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="ffba9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffba9-116">-ResourceGroupName</span></span>
<span data-ttu-id="ffba9-117">Указывает имя группы ресурсов, которой назначена база данных SQL.</span><span class="sxs-lookup"><span data-stu-id="ffba9-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="ffba9-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ffba9-118">-ServerName</span></span>
<span data-ttu-id="ffba9-119">Указывает имя сервера AzureSQL, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="ffba9-119">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="ffba9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffba9-120">-Confirm</span></span>
<span data-ttu-id="ffba9-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ffba9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffba9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffba9-122">-WhatIf</span></span>
<span data-ttu-id="ffba9-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ffba9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffba9-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ffba9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffba9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffba9-125">-DefaultProfile</span></span>
<span data-ttu-id="ffba9-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffba9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffba9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffba9-127">CommonParameters</span></span>
<span data-ttu-id="ffba9-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffba9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffba9-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffba9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffba9-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffba9-130">INPUTS</span></span>

## <span data-ttu-id="ffba9-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffba9-131">OUTPUTS</span></span>

## <span data-ttu-id="ffba9-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffba9-132">NOTES</span></span>

## <span data-ttu-id="ffba9-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffba9-133">RELATED LINKS</span></span>

