---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 07836205ec7311eadf7e48dd79b322d00670f337
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504755"
---
# <span data-ttu-id="d75d3-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d75d3-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="d75d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d75d3-102">SYNOPSIS</span></span>
<span data-ttu-id="d75d3-103">Задает политику геоархивации базы данных.</span><span class="sxs-lookup"><span data-stu-id="d75d3-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="d75d3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d75d3-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d75d3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d75d3-105">DESCRIPTION</span></span>
<span data-ttu-id="d75d3-106">Cmdlet **Set-AzSqlDatabaseGeoBackupPolicy** задает геоархивную политику резервного копирования, зарегистрированную в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d75d3-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="d75d3-107">Это ресурс резервной копии Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="d75d3-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="d75d3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d75d3-108">EXAMPLES</span></span>

## <span data-ttu-id="d75d3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d75d3-109">PARAMETERS</span></span>

### <span data-ttu-id="d75d3-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d75d3-110">-DatabaseName</span></span>
<span data-ttu-id="d75d3-111">Задает имя базы данных, для которой этот cmdlet задает политику геоархивации.</span><span class="sxs-lookup"><span data-stu-id="d75d3-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="d75d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75d3-112">-DefaultProfile</span></span>
<span data-ttu-id="d75d3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d75d3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d75d3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d75d3-114">-ResourceGroupName</span></span>
<span data-ttu-id="d75d3-115">Указывает имя группы ресурсов сервера, который содержит эту базу данных.</span><span class="sxs-lookup"><span data-stu-id="d75d3-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d75d3-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d75d3-116">-ServerName</span></span>
<span data-ttu-id="d75d3-117">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="d75d3-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d75d3-118">-State</span><span class="sxs-lookup"><span data-stu-id="d75d3-118">-State</span></span>
<span data-ttu-id="d75d3-119">Определяет состояние политики геоархивации.</span><span class="sxs-lookup"><span data-stu-id="d75d3-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="d75d3-120">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="d75d3-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d75d3-121">Включено</span><span class="sxs-lookup"><span data-stu-id="d75d3-121">Enabled</span></span> 
- <span data-ttu-id="d75d3-122">Отключено</span><span class="sxs-lookup"><span data-stu-id="d75d3-122">Disabled</span></span>

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

### <span data-ttu-id="d75d3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d75d3-123">-Confirm</span></span>
<span data-ttu-id="d75d3-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75d3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d75d3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d75d3-125">-WhatIf</span></span>
<span data-ttu-id="d75d3-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75d3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d75d3-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d75d3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d75d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75d3-128">CommonParameters</span></span>
<span data-ttu-id="d75d3-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d75d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75d3-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d75d3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75d3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d75d3-131">INPUTS</span></span>

### <span data-ttu-id="d75d3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d75d3-132">System.String</span></span>

## <span data-ttu-id="d75d3-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d75d3-133">OUTPUTS</span></span>

### <span data-ttu-id="d75d3-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d75d3-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="d75d3-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d75d3-135">NOTES</span></span>

## <span data-ttu-id="d75d3-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d75d3-136">RELATED LINKS</span></span>

[<span data-ttu-id="d75d3-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d75d3-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="d75d3-138">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="d75d3-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

