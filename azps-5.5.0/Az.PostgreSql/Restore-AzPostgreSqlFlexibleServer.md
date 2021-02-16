---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: e8554f0ac88cf3d69e36282b7e310cc92b41d6db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213153"
---
# <span data-ttu-id="d0313-101">Restore-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="d0313-101">Restore-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="d0313-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0313-102">SYNOPSIS</span></span>
<span data-ttu-id="d0313-103">Восстановление гибкого сервера PostgreSQL из существующей резервной копии</span><span class="sxs-lookup"><span data-stu-id="d0313-103">Restore a PostgreSQL flexible server from an existing backup</span></span>

## <span data-ttu-id="d0313-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d0313-104">SYNTAX</span></span>

```
Restore-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> -SourceServerName <String>
 -Location <String> -RestorePointInTime <DateTime> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0313-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0313-105">DESCRIPTION</span></span>
<span data-ttu-id="d0313-106">Восстановление сервера из существующей резервной копии</span><span class="sxs-lookup"><span data-stu-id="d0313-106">Restore a server from an existing backup</span></span>

## <span data-ttu-id="d0313-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d0313-107">EXAMPLES</span></span>

### <span data-ttu-id="d0313-108">Пример 1. Восстановление сервера PostgreSql с помощью восстановления PointInTime</span><span class="sxs-lookup"><span data-stu-id="d0313-108">Example 1: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Restore-AzPostgreSqlFlexibleServer -Name pg-restore -ResourceGroupName PowershellPostgreSqlTest -SourceServerName postgresql-test -Location eastus -RestorePointInTime $restorePointInTime 

Name       Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier       
----       -------- ------------------ ------- ----------------------- -------          -------       
pg-restore eastus   postgresql_test         12     131072              Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="d0313-109">Эти cmdlets restore PostgreSql server using PointInTime Restore.</span><span class="sxs-lookup"><span data-stu-id="d0313-109">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="d0313-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0313-110">PARAMETERS</span></span>

### <span data-ttu-id="d0313-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0313-111">-AsJob</span></span>
<span data-ttu-id="d0313-112">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="d0313-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="d0313-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0313-113">-DefaultProfile</span></span>
<span data-ttu-id="d0313-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0313-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0313-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d0313-115">-Location</span></span>
<span data-ttu-id="d0313-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d0313-116">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0313-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d0313-117">-Name</span></span>
<span data-ttu-id="d0313-118">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d0313-118">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0313-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0313-119">-NoWait</span></span>
<span data-ttu-id="d0313-120">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d0313-120">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="d0313-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0313-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0313-122">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d0313-122">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0313-123">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="d0313-123">-RestorePointInTime</span></span>
<span data-ttu-id="d0313-124">Время восстановления (в формате ISO8601), например, 2017-04-26T02:10:00+08:00.</span><span class="sxs-lookup"><span data-stu-id="d0313-124">The point in time to restore from (ISO8601 format), e.g., 2017-04-26T02:10:00+08:00.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0313-125">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="d0313-125">-SourceServerName</span></span>
<span data-ttu-id="d0313-126">Имя сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="d0313-126">The name of the source server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0313-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0313-127">-SubscriptionId</span></span>
<span data-ttu-id="d0313-128">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="d0313-128">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0313-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0313-129">-Confirm</span></span>
<span data-ttu-id="d0313-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d0313-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0313-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0313-131">-WhatIf</span></span>
<span data-ttu-id="d0313-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0313-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0313-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d0313-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0313-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0313-134">CommonParameters</span></span>
<span data-ttu-id="d0313-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0313-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0313-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0313-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0313-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0313-137">INPUTS</span></span>

## <span data-ttu-id="d0313-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d0313-138">OUTPUTS</span></span>

### <span data-ttu-id="d0313-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="d0313-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="d0313-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d0313-140">NOTES</span></span>

<span data-ttu-id="d0313-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d0313-141">ALIASES</span></span>

## <span data-ttu-id="d0313-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0313-142">RELATED LINKS</span></span>

