---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: f1bc8fcc019f25b4337dc88ac55965b8d988e753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566367"
---
# <span data-ttu-id="17bbb-101">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="17bbb-101">Remove-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="17bbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="17bbb-103">Завершает репликацию данных между базой данных SQL и указанной базой данных-получателем.</span><span class="sxs-lookup"><span data-stu-id="17bbb-103">Terminates data replication between a SQL Database and the specified secondary database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17bbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17bbb-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17bbb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="17bbb-106">Командлет **Remove-AzureRmSqlDatabaseSecondary** принудительно прекращает соединение георепликации.</span><span class="sxs-lookup"><span data-stu-id="17bbb-106">The **Remove-AzureRmSqlDatabaseSecondary** cmdlet forces termination of a geo-replication link.</span></span>
<span data-ttu-id="17bbb-107">Этот командлет заменяет командлет Stop-AzureSqlDatabaseCopy.</span><span class="sxs-lookup"><span data-stu-id="17bbb-107">This cmdlet replaces the Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="17bbb-108">Синхронизация репликации перед прекращением работы отсутствует.</span><span class="sxs-lookup"><span data-stu-id="17bbb-108">There is no replication synchronization before termination.</span></span>

## <span data-ttu-id="17bbb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17bbb-109">EXAMPLES</span></span>

## <span data-ttu-id="17bbb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17bbb-110">PARAMETERS</span></span>

### <span data-ttu-id="17bbb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="17bbb-111">-DatabaseName</span></span>
<span data-ttu-id="17bbb-112">Указывает имя основной базы данных SQL Azure с ссылкой репликации, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="17bbb-112">Specifies the name of the primary Azure SQL Database that has the replication link that this cmdlet removes.</span></span>

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

### <span data-ttu-id="17bbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bbb-113">-DefaultProfile</span></span>
<span data-ttu-id="17bbb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="17bbb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17bbb-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17bbb-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="17bbb-116">Указывает имя группы ресурсов для партнеров.</span><span class="sxs-lookup"><span data-stu-id="17bbb-116">Specifies the name of the partner  resource group.</span></span>

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

### <span data-ttu-id="17bbb-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="17bbb-117">-PartnerServerName</span></span>
<span data-ttu-id="17bbb-118">Указывает имя сервера SQL партнера.</span><span class="sxs-lookup"><span data-stu-id="17bbb-118">Specifies the name of the partner SQL Server.</span></span>

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

### <span data-ttu-id="17bbb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17bbb-119">-ResourceGroupName</span></span>
<span data-ttu-id="17bbb-120">Указывает имя группы ресурсов, связанной со ссылкой для репликации, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="17bbb-120">Specifies the name of the resource group that is associated with the replication link to remove.</span></span>

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

### <span data-ttu-id="17bbb-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="17bbb-121">-ServerName</span></span>
<span data-ttu-id="17bbb-122">Указывает имя сервера SQL Server, для которого требуется удалить ссылку для репликации.</span><span class="sxs-lookup"><span data-stu-id="17bbb-122">Specifies the name of the SQL Server that has the replication link to remove.</span></span>

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

### <span data-ttu-id="17bbb-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17bbb-123">-Confirm</span></span>
<span data-ttu-id="17bbb-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17bbb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17bbb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17bbb-125">-WhatIf</span></span>
<span data-ttu-id="17bbb-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17bbb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17bbb-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17bbb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17bbb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bbb-128">CommonParameters</span></span>
<span data-ttu-id="17bbb-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17bbb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bbb-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17bbb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bbb-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17bbb-131">INPUTS</span></span>

### <span data-ttu-id="17bbb-132">System. String</span><span class="sxs-lookup"><span data-stu-id="17bbb-132">System.String</span></span>

## <span data-ttu-id="17bbb-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17bbb-133">OUTPUTS</span></span>

### <span data-ttu-id="17bbb-134">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="17bbb-134">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="17bbb-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="17bbb-135">NOTES</span></span>

## <span data-ttu-id="17bbb-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17bbb-136">RELATED LINKS</span></span>

[<span data-ttu-id="17bbb-137">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="17bbb-137">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="17bbb-138">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="17bbb-138">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="17bbb-139">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="17bbb-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
