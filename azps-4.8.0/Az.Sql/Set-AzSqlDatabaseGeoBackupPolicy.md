---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 07836205ec7311eadf7e48dd79b322d00670f337
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243893"
---
# <span data-ttu-id="f8e58-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f8e58-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="f8e58-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8e58-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e58-103">Задает политику географического резервного копирования базы данных.</span><span class="sxs-lookup"><span data-stu-id="f8e58-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="f8e58-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8e58-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8e58-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8e58-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e58-106">Командлет **Set-AzSqlDatabaseGeoBackupPolicy** задает политику географического резервного копирования, зарегистрированную в базе данных.</span><span class="sxs-lookup"><span data-stu-id="f8e58-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="f8e58-107">Это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="f8e58-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="f8e58-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8e58-108">EXAMPLES</span></span>

## <span data-ttu-id="f8e58-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8e58-109">PARAMETERS</span></span>

### <span data-ttu-id="f8e58-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8e58-110">-DatabaseName</span></span>
<span data-ttu-id="f8e58-111">Указывает имя базы данных, для которой этот командлет задает политику географического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f8e58-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="f8e58-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e58-112">-DefaultProfile</span></span>
<span data-ttu-id="f8e58-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f8e58-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8e58-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e58-114">-ResourceGroupName</span></span>
<span data-ttu-id="f8e58-115">Указывает имя группы ресурсов для сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="f8e58-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="f8e58-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f8e58-116">-ServerName</span></span>
<span data-ttu-id="f8e58-117">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="f8e58-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="f8e58-118">-State</span><span class="sxs-lookup"><span data-stu-id="f8e58-118">-State</span></span>
<span data-ttu-id="f8e58-119">Задает состояние политики географического резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="f8e58-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="f8e58-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f8e58-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8e58-121">Включаем</span><span class="sxs-lookup"><span data-stu-id="f8e58-121">Enabled</span></span> 
- <span data-ttu-id="f8e58-122">Отключает</span><span class="sxs-lookup"><span data-stu-id="f8e58-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e58-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8e58-123">-Confirm</span></span>
<span data-ttu-id="f8e58-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8e58-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8e58-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8e58-125">-WhatIf</span></span>
<span data-ttu-id="f8e58-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8e58-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8e58-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8e58-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8e58-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e58-128">CommonParameters</span></span>
<span data-ttu-id="f8e58-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8e58-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e58-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8e58-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e58-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8e58-131">INPUTS</span></span>

### <span data-ttu-id="f8e58-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f8e58-132">System.String</span></span>

## <span data-ttu-id="f8e58-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8e58-133">OUTPUTS</span></span>

### <span data-ttu-id="f8e58-134">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f8e58-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="f8e58-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8e58-135">NOTES</span></span>

## <span data-ttu-id="f8e58-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8e58-136">RELATED LINKS</span></span>

[<span data-ttu-id="f8e58-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="f8e58-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="f8e58-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f8e58-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
