---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077556"
---
# <span data-ttu-id="2f5d9-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="2f5d9-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="2f5d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="2f5d9-103">Создание ключа агента синхронизации SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="2f5d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f5d9-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f5d9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f5d9-105">DESCRIPTION</span></span>
<span data-ttu-id="2f5d9-106">Командлет **New-AzSqlSyncAgentKey** создает ключ агента синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="2f5d9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f5d9-107">EXAMPLES</span></span>

### <span data-ttu-id="2f5d9-108">Пример 1: создание ключа агента синхронизации для агента синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="2f5d9-109">Эта команда создает ключ агента синхронизации для агента Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="2f5d9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f5d9-110">PARAMETERS</span></span>

### <span data-ttu-id="2f5d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f5d9-111">-DefaultProfile</span></span>
<span data-ttu-id="2f5d9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2f5d9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f5d9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f5d9-113">-ResourceGroupName</span></span>
<span data-ttu-id="2f5d9-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="2f5d9-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2f5d9-115">-ServerName</span></span>
<span data-ttu-id="2f5d9-116">Имя сервера Azure SQL Server, в котором находится агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="2f5d9-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="2f5d9-117">-SyncAgentName</span></span>
<span data-ttu-id="2f5d9-118">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-118">The sync agent name.</span></span>

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

### <span data-ttu-id="2f5d9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f5d9-119">-Confirm</span></span>
<span data-ttu-id="2f5d9-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f5d9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f5d9-121">-WhatIf</span></span>
<span data-ttu-id="2f5d9-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f5d9-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f5d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f5d9-124">CommonParameters</span></span>
<span data-ttu-id="2f5d9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f5d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f5d9-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f5d9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f5d9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f5d9-127">INPUTS</span></span>

### <span data-ttu-id="2f5d9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2f5d9-128">System.String</span></span>

## <span data-ttu-id="2f5d9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f5d9-129">OUTPUTS</span></span>

### <span data-ttu-id="2f5d9-130">Microsoft. Azure. Commands. SQL. Sync. Model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="2f5d9-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="2f5d9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f5d9-131">NOTES</span></span>

## <span data-ttu-id="2f5d9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f5d9-132">RELATED LINKS</span></span>
