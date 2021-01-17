---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417767"
---
# <span data-ttu-id="2ecb7-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2ecb7-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="2ecb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ecb7-102">SYNOPSIS</span></span>
<span data-ttu-id="2ecb7-103">Подробные сведения о сопоставлении контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="2ecb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ecb7-104">SYNTAX</span></span>

### <span data-ttu-id="2ecb7-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ecb7-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ecb7-106">Получить</span><span class="sxs-lookup"><span data-stu-id="2ecb7-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2ecb7-107">Список</span><span class="sxs-lookup"><span data-stu-id="2ecb7-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ecb7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ecb7-108">DESCRIPTION</span></span>
<span data-ttu-id="2ecb7-109">Подробные сведения о сопоставлении контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="2ecb7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ecb7-110">EXAMPLES</span></span>

### <span data-ttu-id="2ecb7-111">Пример 1. Сопоставление</span><span class="sxs-lookup"><span data-stu-id="2ecb7-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="2ecb7-112">Получите подробные подробности о сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-112">Get a mapping detail.</span></span>

## <span data-ttu-id="2ecb7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ecb7-113">PARAMETERS</span></span>

### <span data-ttu-id="2ecb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ecb7-114">-DefaultProfile</span></span>
<span data-ttu-id="2ecb7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ecb7-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="2ecb7-116">-FabricName</span></span>
<span data-ttu-id="2ecb7-117">Имя ткань.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-117">Fabric name.</span></span>

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

### <span data-ttu-id="2ecb7-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="2ecb7-118">-MappingName</span></span>
<span data-ttu-id="2ecb7-119">Имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="2ecb7-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="2ecb7-120">-ProtectionContainerName</span></span>
<span data-ttu-id="2ecb7-121">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-121">Protection container name.</span></span>

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

### <span data-ttu-id="2ecb7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ecb7-122">-ResourceGroupName</span></span>
<span data-ttu-id="2ecb7-123">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="2ecb7-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2ecb7-124">-ResourceName</span></span>
<span data-ttu-id="2ecb7-125">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="2ecb7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ecb7-126">-SubscriptionId</span></span>
<span data-ttu-id="2ecb7-127">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-127">The subscription Id.</span></span>

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

### <span data-ttu-id="2ecb7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ecb7-128">CommonParameters</span></span>
<span data-ttu-id="2ecb7-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ecb7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ecb7-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ecb7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ecb7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ecb7-131">INPUTS</span></span>

## <span data-ttu-id="2ecb7-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ecb7-132">OUTPUTS</span></span>

### <span data-ttu-id="2ecb7-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2ecb7-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="2ecb7-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ecb7-134">NOTES</span></span>

<span data-ttu-id="2ecb7-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2ecb7-135">ALIASES</span></span>

## <span data-ttu-id="2ecb7-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ecb7-136">RELATED LINKS</span></span>

