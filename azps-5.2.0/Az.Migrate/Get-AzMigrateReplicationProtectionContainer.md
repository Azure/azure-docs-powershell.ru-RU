---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328120"
---
# <span data-ttu-id="a5b37-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a5b37-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="a5b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b37-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b37-103">Сведения о контейнере защиты.</span><span class="sxs-lookup"><span data-stu-id="a5b37-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="a5b37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5b37-104">SYNTAX</span></span>

### <span data-ttu-id="a5b37-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5b37-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a5b37-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a5b37-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5b37-107">Список1</span><span class="sxs-lookup"><span data-stu-id="a5b37-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a5b37-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b37-108">DESCRIPTION</span></span>
<span data-ttu-id="a5b37-109">Сведения о контейнере защиты.</span><span class="sxs-lookup"><span data-stu-id="a5b37-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="a5b37-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5b37-110">EXAMPLES</span></span>

### <span data-ttu-id="a5b37-111">Пример 1. Список всех контейнеров защиты в хранилище и ткань</span><span class="sxs-lookup"><span data-stu-id="a5b37-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="a5b37-112">Все списки.</span><span class="sxs-lookup"><span data-stu-id="a5b37-112">Lists all.</span></span>

### <span data-ttu-id="a5b37-113">Пример 2. Получить определенный контейнер</span><span class="sxs-lookup"><span data-stu-id="a5b37-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="a5b37-114">Возвращает конкретное.</span><span class="sxs-lookup"><span data-stu-id="a5b37-114">Gets a specific one.</span></span>

## <span data-ttu-id="a5b37-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5b37-115">PARAMETERS</span></span>

### <span data-ttu-id="a5b37-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b37-116">-DefaultProfile</span></span>
<span data-ttu-id="a5b37-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b37-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b37-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="a5b37-118">-FabricName</span></span>
<span data-ttu-id="a5b37-119">Имя ткань.</span><span class="sxs-lookup"><span data-stu-id="a5b37-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b37-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="a5b37-120">-ProtectionContainerName</span></span>
<span data-ttu-id="a5b37-121">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="a5b37-121">Protection container name.</span></span>

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

### <span data-ttu-id="a5b37-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b37-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5b37-123">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a5b37-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="a5b37-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a5b37-124">-ResourceName</span></span>
<span data-ttu-id="a5b37-125">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a5b37-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="a5b37-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5b37-126">-SubscriptionId</span></span>
<span data-ttu-id="a5b37-127">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="a5b37-127">The subscription Id.</span></span>

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

### <span data-ttu-id="a5b37-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b37-128">CommonParameters</span></span>
<span data-ttu-id="a5b37-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b37-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b37-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5b37-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b37-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5b37-131">INPUTS</span></span>

## <span data-ttu-id="a5b37-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5b37-132">OUTPUTS</span></span>

### <span data-ttu-id="a5b37-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a5b37-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="a5b37-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5b37-134">NOTES</span></span>

<span data-ttu-id="a5b37-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a5b37-135">ALIASES</span></span>

## <span data-ttu-id="a5b37-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5b37-136">RELATED LINKS</span></span>

