---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 9ffccf1122ac9919758883100eacce7933f5fea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562059"
---
# <span data-ttu-id="716bc-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="716bc-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="716bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="716bc-102">SYNOPSIS</span></span>
<span data-ttu-id="716bc-103">Получает удаленную базу данных, которую можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="716bc-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="716bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="716bc-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="716bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="716bc-105">DESCRIPTION</span></span>
<span data-ttu-id="716bc-106">Командлет **Get-AzureRMSqlDeletedDatabaseBackup** возвращает указанное удаленное резервное копирование базы данных SQL, которое можно восстановить, или все удаленные резервные копии, которые можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="716bc-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="716bc-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="716bc-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="716bc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="716bc-108">EXAMPLES</span></span>

### <span data-ttu-id="716bc-109">Пример 1: получение всех удаленных резервных копий базы данных на сервере</span><span class="sxs-lookup"><span data-stu-id="716bc-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="716bc-110">Эта команда возвращает все удаленные резервные копии базы данных на сервере.</span><span class="sxs-lookup"><span data-stu-id="716bc-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="716bc-111">Пример 2: получение указанной удаленной резервной копии базы данных</span><span class="sxs-lookup"><span data-stu-id="716bc-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="716bc-112">Эта команда возвращает удаленное резервное копирование базы данных для ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="716bc-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="716bc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="716bc-113">PARAMETERS</span></span>

### <span data-ttu-id="716bc-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="716bc-114">-DatabaseName</span></span>
<span data-ttu-id="716bc-115">Указывает имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="716bc-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="716bc-116">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="716bc-116">-DeletionDate</span></span>
<span data-ttu-id="716bc-117">Указывает дату удаления базы данных в виде объекта **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="716bc-117">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="716bc-118">Чтобы получить объект **DateTime** , используйте командлет Get-Date.</span><span class="sxs-lookup"><span data-stu-id="716bc-118">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="716bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="716bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="716bc-120">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="716bc-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="716bc-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="716bc-121">-ServerName</span></span>
<span data-ttu-id="716bc-122">Указывает имя сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="716bc-122">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="716bc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="716bc-123">-Confirm</span></span>
<span data-ttu-id="716bc-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="716bc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="716bc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="716bc-125">-WhatIf</span></span>
<span data-ttu-id="716bc-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="716bc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="716bc-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="716bc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="716bc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="716bc-128">-DefaultProfile</span></span>
<span data-ttu-id="716bc-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="716bc-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="716bc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="716bc-130">CommonParameters</span></span>
<span data-ttu-id="716bc-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="716bc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="716bc-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="716bc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="716bc-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="716bc-133">INPUTS</span></span>

## <span data-ttu-id="716bc-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="716bc-134">OUTPUTS</span></span>

## <span data-ttu-id="716bc-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="716bc-135">NOTES</span></span>

## <span data-ttu-id="716bc-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="716bc-136">RELATED LINKS</span></span>

[<span data-ttu-id="716bc-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="716bc-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="716bc-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="716bc-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
