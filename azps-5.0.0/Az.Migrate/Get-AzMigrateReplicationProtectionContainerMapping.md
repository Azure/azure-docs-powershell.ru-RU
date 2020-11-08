---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250064"
---
# <span data-ttu-id="56739-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="56739-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="56739-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56739-102">SYNOPSIS</span></span>
<span data-ttu-id="56739-103">Получает сведения о сопоставлении контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="56739-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="56739-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56739-104">SYNTAX</span></span>

### <span data-ttu-id="56739-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56739-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56739-106">Получить</span><span class="sxs-lookup"><span data-stu-id="56739-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56739-107">Список</span><span class="sxs-lookup"><span data-stu-id="56739-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="56739-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56739-108">DESCRIPTION</span></span>
<span data-ttu-id="56739-109">Получает сведения о сопоставлении контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="56739-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="56739-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56739-110">EXAMPLES</span></span>

### <span data-ttu-id="56739-111">Пример 1: получение определенного сопоставления</span><span class="sxs-lookup"><span data-stu-id="56739-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="56739-112">Получение сведений о сопоставлении.</span><span class="sxs-lookup"><span data-stu-id="56739-112">Get a mapping detail.</span></span>

## <span data-ttu-id="56739-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56739-113">PARAMETERS</span></span>

### <span data-ttu-id="56739-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56739-114">-DefaultProfile</span></span>
<span data-ttu-id="56739-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56739-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56739-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="56739-116">-FabricName</span></span>
<span data-ttu-id="56739-117">Имя структуры.</span><span class="sxs-lookup"><span data-stu-id="56739-117">Fabric name.</span></span>

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

### <span data-ttu-id="56739-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="56739-118">-MappingName</span></span>
<span data-ttu-id="56739-119">Имя сопоставления контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="56739-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="56739-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="56739-120">-ProtectionContainerName</span></span>
<span data-ttu-id="56739-121">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="56739-121">Protection container name.</span></span>

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

### <span data-ttu-id="56739-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56739-122">-ResourceGroupName</span></span>
<span data-ttu-id="56739-123">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="56739-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="56739-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="56739-124">-ResourceName</span></span>
<span data-ttu-id="56739-125">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="56739-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="56739-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56739-126">-SubscriptionId</span></span>
<span data-ttu-id="56739-127">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="56739-127">The subscription Id.</span></span>

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

### <span data-ttu-id="56739-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56739-128">CommonParameters</span></span>
<span data-ttu-id="56739-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56739-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56739-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56739-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56739-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56739-131">INPUTS</span></span>

## <span data-ttu-id="56739-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56739-132">OUTPUTS</span></span>

### <span data-ttu-id="56739-133">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="56739-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="56739-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="56739-134">NOTES</span></span>

<span data-ttu-id="56739-135">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="56739-135">ALIASES</span></span>

## <span data-ttu-id="56739-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56739-136">RELATED LINKS</span></span>

