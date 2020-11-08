---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250067"
---
# <span data-ttu-id="671fd-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="671fd-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="671fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="671fd-102">SYNOPSIS</span></span>
<span data-ttu-id="671fd-103">Получает сведения о контейнере защиты.</span><span class="sxs-lookup"><span data-stu-id="671fd-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="671fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="671fd-104">SYNTAX</span></span>

### <span data-ttu-id="671fd-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="671fd-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="671fd-106">Получить</span><span class="sxs-lookup"><span data-stu-id="671fd-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="671fd-107">List1</span><span class="sxs-lookup"><span data-stu-id="671fd-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="671fd-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="671fd-108">DESCRIPTION</span></span>
<span data-ttu-id="671fd-109">Получает сведения о контейнере защиты.</span><span class="sxs-lookup"><span data-stu-id="671fd-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="671fd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="671fd-110">EXAMPLES</span></span>

### <span data-ttu-id="671fd-111">Пример 1: список всех контейнеров защиты в хранилище и структуре</span><span class="sxs-lookup"><span data-stu-id="671fd-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="671fd-112">Список всех.</span><span class="sxs-lookup"><span data-stu-id="671fd-112">Lists all.</span></span>

### <span data-ttu-id="671fd-113">Пример 2: получение определенного контейнера</span><span class="sxs-lookup"><span data-stu-id="671fd-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="671fd-114">Возвращает определенный элемент.</span><span class="sxs-lookup"><span data-stu-id="671fd-114">Gets a specific one.</span></span>

## <span data-ttu-id="671fd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="671fd-115">PARAMETERS</span></span>

### <span data-ttu-id="671fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="671fd-116">-DefaultProfile</span></span>
<span data-ttu-id="671fd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="671fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="671fd-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="671fd-118">-FabricName</span></span>
<span data-ttu-id="671fd-119">Имя структуры.</span><span class="sxs-lookup"><span data-stu-id="671fd-119">Fabric name.</span></span>

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

### <span data-ttu-id="671fd-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="671fd-120">-ProtectionContainerName</span></span>
<span data-ttu-id="671fd-121">Имя контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="671fd-121">Protection container name.</span></span>

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

### <span data-ttu-id="671fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="671fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="671fd-123">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="671fd-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="671fd-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="671fd-124">-ResourceName</span></span>
<span data-ttu-id="671fd-125">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="671fd-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="671fd-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="671fd-126">-SubscriptionId</span></span>
<span data-ttu-id="671fd-127">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="671fd-127">The subscription Id.</span></span>

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

### <span data-ttu-id="671fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="671fd-128">CommonParameters</span></span>
<span data-ttu-id="671fd-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="671fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="671fd-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="671fd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="671fd-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="671fd-131">INPUTS</span></span>

## <span data-ttu-id="671fd-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="671fd-132">OUTPUTS</span></span>

### <span data-ttu-id="671fd-133">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="671fd-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="671fd-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="671fd-134">NOTES</span></span>

<span data-ttu-id="671fd-135">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="671fd-135">ALIASES</span></span>

## <span data-ttu-id="671fd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="671fd-136">RELATED LINKS</span></span>

