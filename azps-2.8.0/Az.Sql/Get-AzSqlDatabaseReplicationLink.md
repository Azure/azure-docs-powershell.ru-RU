---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 40054224-52FF-4AF6-A090-9F6D07A2BA99
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasereplicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseReplicationLink.md
ms.openlocfilehash: 6bb2a3891abe8453ee8460f6879dbc134f6ab29b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906226"
---
# <span data-ttu-id="3caff-101">Get-AzSqlDatabaseReplicationLink</span><span class="sxs-lookup"><span data-stu-id="3caff-101">Get-AzSqlDatabaseReplicationLink</span></span>

## <span data-ttu-id="3caff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3caff-102">SYNOPSIS</span></span>
<span data-ttu-id="3caff-103">Получает ссылки георепликации между базой данных Azure SQL и группой ресурсов или SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3caff-103">Gets the geo-replication links between an Azure SQL Database and a resource group or SQL Server.</span></span>

## <span data-ttu-id="3caff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3caff-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseReplicationLink [-DatabaseName] <String> -PartnerResourceGroupName <String>
 [-PartnerServerName <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3caff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3caff-105">DESCRIPTION</span></span>
<span data-ttu-id="3caff-106">Командлет **Get-AzSqlDatabaseReplicationLink** заменяет командлет **Get-AzSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="3caff-106">The **Get-AzSqlDatabaseReplicationLink** cmdlet replaces the **Get-AzSqlDatabaseCopy** cmdlet.</span></span>
<span data-ttu-id="3caff-107">Она получает все ссылки георепликации между указанной базой данных Azure SQL и группой ресурсов или сервером AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="3caff-107">It gets all geo-replication links between the specified Azure SQL Database and a resource group or AzureSQL Server.</span></span>

## <span data-ttu-id="3caff-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3caff-108">EXAMPLES</span></span>

## <span data-ttu-id="3caff-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3caff-109">PARAMETERS</span></span>

### <span data-ttu-id="3caff-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3caff-110">-DatabaseName</span></span>
<span data-ttu-id="3caff-111">Указывает имя базы данных SQL, для которой требуется получить ссылки.</span><span class="sxs-lookup"><span data-stu-id="3caff-111">Specifies the name of the SQL Database for which to retrieve links.</span></span>

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

### <span data-ttu-id="3caff-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3caff-112">-DefaultProfile</span></span>
<span data-ttu-id="3caff-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3caff-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3caff-114">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3caff-114">-PartnerResourceGroupName</span></span>
<span data-ttu-id="3caff-115">Указывает имя группы ресурсов, которой назначен партнер.</span><span class="sxs-lookup"><span data-stu-id="3caff-115">Specifies the name of the resource group to which the partner is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3caff-116">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="3caff-116">-PartnerServerName</span></span>
<span data-ttu-id="3caff-117">Указывает имя сервера Azure SQL Server для партнера.</span><span class="sxs-lookup"><span data-stu-id="3caff-117">Specifies the name of the Azure SQL Server for the partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="3caff-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3caff-118">-ResourceGroupName</span></span>
<span data-ttu-id="3caff-119">Указывает имя группы ресурсов Azure для базы данных, для которой требуется получить ссылки.</span><span class="sxs-lookup"><span data-stu-id="3caff-119">Specifies the name of the Azure resource group for the database for which to retrieve links.</span></span>

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

### <span data-ttu-id="3caff-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3caff-120">-ServerName</span></span>
<span data-ttu-id="3caff-121">Указывает имя сервера SQL Server для базы данных, для которого требуется получить ссылки.</span><span class="sxs-lookup"><span data-stu-id="3caff-121">Specifies the name of the SQL Server for the database to retrieve links for.</span></span>

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

### <span data-ttu-id="3caff-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3caff-122">-Confirm</span></span>
<span data-ttu-id="3caff-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3caff-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3caff-124">-WhatIf</span></span>
<span data-ttu-id="3caff-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3caff-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3caff-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3caff-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3caff-127">CommonParameters</span></span>
<span data-ttu-id="3caff-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3caff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3caff-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3caff-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3caff-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3caff-130">INPUTS</span></span>

### <span data-ttu-id="3caff-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3caff-131">System.String</span></span>

## <span data-ttu-id="3caff-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3caff-132">OUTPUTS</span></span>

### <span data-ttu-id="3caff-133">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="3caff-133">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="3caff-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="3caff-134">NOTES</span></span>

## <span data-ttu-id="3caff-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3caff-135">RELATED LINKS</span></span>

[<span data-ttu-id="3caff-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3caff-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
