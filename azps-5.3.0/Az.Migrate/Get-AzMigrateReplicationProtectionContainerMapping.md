---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505089"
---
# <span data-ttu-id="e2cac-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e2cac-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="e2cac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2cac-102">SYNOPSIS</span></span>
<span data-ttu-id="e2cac-103">Подробные сведения о сопоставлении контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="e2cac-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="e2cac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e2cac-104">SYNTAX</span></span>

### <span data-ttu-id="e2cac-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e2cac-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e2cac-106">Получить</span><span class="sxs-lookup"><span data-stu-id="e2cac-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e2cac-107">Список</span><span class="sxs-lookup"><span data-stu-id="e2cac-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2cac-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e2cac-108">DESCRIPTION</span></span>
<span data-ttu-id="e2cac-109">Подробные сведения о сопоставлении контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="e2cac-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="e2cac-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e2cac-110">EXAMPLES</span></span>

### <span data-ttu-id="e2cac-111">Пример 1. Сопоставление</span><span class="sxs-lookup"><span data-stu-id="e2cac-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="e2cac-112">Получите подробные подробности о сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="e2cac-112">Get a mapping detail.</span></span>

## <span data-ttu-id="e2cac-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2cac-113">PARAMETERS</span></span>

### <span data-ttu-id="e2cac-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2cac-114">-DefaultProfile</span></span>
<span data-ttu-id="e2cac-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e2cac-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2cac-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="e2cac-116">-FabricName</span></span>
<span data-ttu-id="e2cac-117">Имя ткань.</span><span class="sxs-lookup"><span data-stu-id="e2cac-117">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2cac-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="e2cac-118">-MappingName</span></span>
<span data-ttu-id="e2cac-119">Имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="e2cac-119">Protection Container mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2cac-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="e2cac-120">-ProtectionContainerName</span></span>
<span data-ttu-id="e2cac-121">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="e2cac-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2cac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2cac-122">-ResourceGroupName</span></span>
<span data-ttu-id="e2cac-123">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2cac-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="e2cac-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e2cac-124">-ResourceName</span></span>
<span data-ttu-id="e2cac-125">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e2cac-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="e2cac-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2cac-126">-SubscriptionId</span></span>
<span data-ttu-id="e2cac-127">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="e2cac-127">The subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2cac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2cac-128">CommonParameters</span></span>
<span data-ttu-id="e2cac-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2cac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2cac-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2cac-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2cac-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2cac-131">INPUTS</span></span>

## <span data-ttu-id="e2cac-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2cac-132">OUTPUTS</span></span>

### <span data-ttu-id="e2cac-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e2cac-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="e2cac-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e2cac-134">NOTES</span></span>

<span data-ttu-id="e2cac-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e2cac-135">ALIASES</span></span>

## <span data-ttu-id="e2cac-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e2cac-136">RELATED LINKS</span></span>

