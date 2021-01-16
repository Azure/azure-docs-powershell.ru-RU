---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncAgentKey.md
ms.openlocfilehash: e6ccf84d2de6c64000a6663de5a5b696d9033eae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394967"
---
# <span data-ttu-id="82acd-101">New-AzSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="82acd-101">New-AzSqlSyncAgentKey</span></span>

## <span data-ttu-id="82acd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82acd-102">SYNOPSIS</span></span>
<span data-ttu-id="82acd-103">Создает ключ агента синхронизации SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="82acd-103">Creates an Azure SQL Sync Agent Key.</span></span>

## <span data-ttu-id="82acd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82acd-104">SYNTAX</span></span>

```
New-AzSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82acd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82acd-105">DESCRIPTION</span></span>
<span data-ttu-id="82acd-106">Для создания ключа агента синхронизации Azure SQL **AzSqlSyncAgentKey.**</span><span class="sxs-lookup"><span data-stu-id="82acd-106">The **New-AzSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="82acd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82acd-107">EXAMPLES</span></span>

### <span data-ttu-id="82acd-108">Пример 1. Создание ключа агента синхронизации для агента синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="82acd-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="82acd-109">Эта команда создает ключ агента синхронизации для azure SQL синхронизации.</span><span class="sxs-lookup"><span data-stu-id="82acd-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="82acd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82acd-110">PARAMETERS</span></span>

### <span data-ttu-id="82acd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82acd-111">-DefaultProfile</span></span>
<span data-ttu-id="82acd-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82acd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82acd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82acd-113">-ResourceGroupName</span></span>
<span data-ttu-id="82acd-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="82acd-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="82acd-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="82acd-115">-ServerName</span></span>
<span data-ttu-id="82acd-116">Имя Azure, SQL Server агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="82acd-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="82acd-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="82acd-117">-SyncAgentName</span></span>
<span data-ttu-id="82acd-118">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="82acd-118">The sync agent name.</span></span>

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

### <span data-ttu-id="82acd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82acd-119">-Confirm</span></span>
<span data-ttu-id="82acd-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82acd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82acd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82acd-121">-WhatIf</span></span>
<span data-ttu-id="82acd-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82acd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82acd-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82acd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82acd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82acd-124">CommonParameters</span></span>
<span data-ttu-id="82acd-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82acd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82acd-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82acd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82acd-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82acd-127">INPUTS</span></span>

### <span data-ttu-id="82acd-128">System.String</span><span class="sxs-lookup"><span data-stu-id="82acd-128">System.String</span></span>

## <span data-ttu-id="82acd-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82acd-129">OUTPUTS</span></span>

### <span data-ttu-id="82acd-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="82acd-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="82acd-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82acd-131">NOTES</span></span>

## <span data-ttu-id="82acd-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82acd-132">RELATED LINKS</span></span>
