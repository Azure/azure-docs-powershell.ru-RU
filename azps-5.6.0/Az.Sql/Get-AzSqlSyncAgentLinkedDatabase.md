---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: b27aee4c665dd2725bfd8643cb12ca005a5c4e1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014499"
---
# <span data-ttu-id="1fa07-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="1fa07-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="1fa07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fa07-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa07-103">Возвращает сведения о базах SQL Server, связанных агентом синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1fa07-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="1fa07-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1fa07-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fa07-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fa07-105">DESCRIPTION</span></span>
<span data-ttu-id="1fa07-106">Cmdlet **Get-AzSqlSyncAgentLinkedDatabase** возвращает сведения о базе SQL Server, связанных агентом синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1fa07-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="1fa07-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1fa07-107">EXAMPLES</span></span>

### <span data-ttu-id="1fa07-108">Пример 1. Получите связанные базы SQL Server для агента синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1fa07-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="1fa07-109">В следующем примере возвращаются связанные SQL Server базы данных, связанные агентом синхронизации Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1fa07-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="1fa07-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fa07-110">PARAMETERS</span></span>

### <span data-ttu-id="1fa07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fa07-111">-DefaultProfile</span></span>
<span data-ttu-id="1fa07-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1fa07-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fa07-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fa07-113">-ResourceGroupName</span></span>
<span data-ttu-id="1fa07-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fa07-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="1fa07-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1fa07-115">-ServerName</span></span>
<span data-ttu-id="1fa07-116">Имя Azure, SQL Server агент синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1fa07-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="1fa07-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="1fa07-117">-SyncAgentName</span></span>
<span data-ttu-id="1fa07-118">Имя агента синхронизации.</span><span class="sxs-lookup"><span data-stu-id="1fa07-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fa07-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa07-119">CommonParameters</span></span>
<span data-ttu-id="1fa07-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fa07-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa07-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fa07-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa07-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fa07-122">INPUTS</span></span>

### <span data-ttu-id="1fa07-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1fa07-123">System.String</span></span>

## <span data-ttu-id="1fa07-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1fa07-124">OUTPUTS</span></span>

### <span data-ttu-id="1fa07-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1fa07-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="1fa07-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1fa07-126">NOTES</span></span>

## <span data-ttu-id="1fa07-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fa07-127">RELATED LINKS</span></span>
