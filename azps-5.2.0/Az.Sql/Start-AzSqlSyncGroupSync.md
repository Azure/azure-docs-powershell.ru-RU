---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqlsyncgroupsync
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlSyncGroupSync.md
ms.openlocfilehash: e35187bf22015f3398a9fd95ce60a1cd597f7c22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400748"
---
# <span data-ttu-id="a2c36-101">Start-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a2c36-101">Start-AzSqlSyncGroupSync</span></span>

## <span data-ttu-id="a2c36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c36-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c36-103">Запускает синхронизацию группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a2c36-103">Starts a sync group synchronization.</span></span>

## <span data-ttu-id="a2c36-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a2c36-104">SYNTAX</span></span>

```
Start-AzSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2c36-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2c36-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c36-106">Для начала синхронизации группы синхронизации запускается команда **Start-AzSqlSyncGroupSync.**</span><span class="sxs-lookup"><span data-stu-id="a2c36-106">The **Start-AzSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="a2c36-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a2c36-107">EXAMPLES</span></span>

### <span data-ttu-id="a2c36-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2c36-108">Example 1</span></span>
```
PS C:\> Start-AzSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="a2c36-109">Эта команда запускает этап синхронизации для mysg группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a2c36-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="a2c36-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2c36-110">PARAMETERS</span></span>

### <span data-ttu-id="a2c36-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2c36-111">-DatabaseName</span></span>
<span data-ttu-id="a2c36-112">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a2c36-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="a2c36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c36-113">-DefaultProfile</span></span>
<span data-ttu-id="a2c36-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a2c36-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2c36-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2c36-115">-PassThru</span></span>
<span data-ttu-id="a2c36-116">Определяет, возвращает ли группа синхронизации</span><span class="sxs-lookup"><span data-stu-id="a2c36-116">Defines Whether return the sync group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c36-117">-ResourceGroupName</span></span>
<span data-ttu-id="a2c36-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a2c36-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="a2c36-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a2c36-119">-ServerName</span></span>
<span data-ttu-id="a2c36-120">Имя службы Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a2c36-120">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="a2c36-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c36-121">-SyncGroupName</span></span>
<span data-ttu-id="a2c36-122">Имя группы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="a2c36-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2c36-123">-Confirm</span></span>
<span data-ttu-id="a2c36-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a2c36-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2c36-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c36-125">-WhatIf</span></span>
<span data-ttu-id="a2c36-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2c36-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c36-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a2c36-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2c36-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c36-128">CommonParameters</span></span>
<span data-ttu-id="a2c36-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2c36-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c36-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2c36-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c36-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2c36-131">INPUTS</span></span>

### <span data-ttu-id="a2c36-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a2c36-132">System.String</span></span>

## <span data-ttu-id="a2c36-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a2c36-133">OUTPUTS</span></span>

### <span data-ttu-id="a2c36-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="a2c36-134">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="a2c36-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a2c36-135">NOTES</span></span>

## <span data-ttu-id="a2c36-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2c36-136">RELATED LINKS</span></span>

[<span data-ttu-id="a2c36-137">Stop-AzSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="a2c36-137">Stop-AzSqlSyncGroupSync</span></span>](./Stop-AzSqlSyncGroupSync.md)

