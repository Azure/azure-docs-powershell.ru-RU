---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 4353a61efd0141947879ad6795c321f5ed43e1d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235794"
---
# <span data-ttu-id="f6935-101">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f6935-101">Remove-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="f6935-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6935-102">SYNOPSIS</span></span>
<span data-ttu-id="f6935-103">Завершает репликацию данных между базой данных SQL и указанной базой данных-получателем.</span><span class="sxs-lookup"><span data-stu-id="f6935-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

## <span data-ttu-id="f6935-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6935-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6935-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6935-105">DESCRIPTION</span></span>
<span data-ttu-id="f6935-106">Командлет **Remove-AzSqlDatabaseSecondary** принудительно прекращает соединение георепликации.</span><span class="sxs-lookup"><span data-stu-id="f6935-106">The **Remove-AzSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="f6935-107">Этот командлет заменяет командлет Stop-AzSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="f6935-107">This cmdlet replaces the Stop-AzSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="f6935-108">Синхронизация репликации перед прекращением работы отсутствует.</span><span class="sxs-lookup"><span data-stu-id="f6935-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="f6935-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6935-109">EXAMPLES</span></span>

## <span data-ttu-id="f6935-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6935-110">PARAMETERS</span></span>

### <span data-ttu-id="f6935-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6935-111">-DatabaseName</span></span>
<span data-ttu-id="f6935-112">Указывает имя основной базы данных SQL Azure с ссылкой репликации, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f6935-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f6935-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6935-113">-DefaultProfile</span></span>
<span data-ttu-id="f6935-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f6935-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6935-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6935-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f6935-116">Указывает имя группы ресурсов для партнеров.</span><span class="sxs-lookup"><span data-stu-id="f6935-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="f6935-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="f6935-117">-PartnerServerName</span></span>
<span data-ttu-id="f6935-118">Указывает имя сервера SQL партнера.</span><span class="sxs-lookup"><span data-stu-id="f6935-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="f6935-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6935-119">-ResourceGroupName</span></span>
<span data-ttu-id="f6935-120">Указывает имя группы ресурсов, связанной со ссылкой для репликации, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f6935-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="f6935-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f6935-121">-ServerName</span></span>
<span data-ttu-id="f6935-122">Указывает имя сервера SQL Server, для которого требуется удалить ссылку для репликации.</span><span class="sxs-lookup"><span data-stu-id="f6935-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="f6935-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6935-123">-Confirm</span></span>
<span data-ttu-id="f6935-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6935-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6935-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6935-125">-WhatIf</span></span>
<span data-ttu-id="f6935-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6935-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6935-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6935-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6935-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6935-128">CommonParameters</span></span>
<span data-ttu-id="f6935-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6935-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6935-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6935-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6935-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6935-131">INPUTS</span></span>

### <span data-ttu-id="f6935-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f6935-132">System.String</span></span>

## <span data-ttu-id="f6935-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6935-133">OUTPUTS</span></span>

### <span data-ttu-id="f6935-134">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="f6935-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="f6935-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6935-135">NOTES</span></span>

## <span data-ttu-id="f6935-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6935-136">RELATED LINKS</span></span>

[<span data-ttu-id="f6935-137">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f6935-137">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f6935-138">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f6935-138">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f6935-139">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f6935-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
