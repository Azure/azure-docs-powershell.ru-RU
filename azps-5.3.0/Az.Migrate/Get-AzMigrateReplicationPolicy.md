---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518242"
---
# <span data-ttu-id="0a5d9-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="0a5d9-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="0a5d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5d9-103">Возвращает сведения о политике репликации.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="0a5d9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a5d9-104">SYNTAX</span></span>

### <span data-ttu-id="0a5d9-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a5d9-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a5d9-106">Получить</span><span class="sxs-lookup"><span data-stu-id="0a5d9-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0a5d9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a5d9-107">DESCRIPTION</span></span>
<span data-ttu-id="0a5d9-108">Возвращает сведения о политике репликации.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="0a5d9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a5d9-109">EXAMPLES</span></span>

### <span data-ttu-id="0a5d9-110">Пример 1. Все политики в хранилище</span><span class="sxs-lookup"><span data-stu-id="0a5d9-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="0a5d9-111">Получите все политики.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-111">Get all policies.</span></span>

### <span data-ttu-id="0a5d9-112">Пример 2. Получить определенную политику</span><span class="sxs-lookup"><span data-stu-id="0a5d9-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="0a5d9-113">Получите конкретный.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-113">Get a specific one.</span></span>

## <span data-ttu-id="0a5d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a5d9-114">PARAMETERS</span></span>

### <span data-ttu-id="0a5d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5d9-115">-DefaultProfile</span></span>
<span data-ttu-id="0a5d9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a5d9-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="0a5d9-117">-PolicyName</span></span>
<span data-ttu-id="0a5d9-118">Имя политики репликации.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-118">Replication policy name.</span></span>

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

### <span data-ttu-id="0a5d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a5d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="0a5d9-120">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="0a5d9-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0a5d9-121">-ResourceName</span></span>
<span data-ttu-id="0a5d9-122">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="0a5d9-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a5d9-123">-SubscriptionId</span></span>
<span data-ttu-id="0a5d9-124">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-124">The subscription Id.</span></span>

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

### <span data-ttu-id="0a5d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5d9-125">CommonParameters</span></span>
<span data-ttu-id="0a5d9-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a5d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5d9-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a5d9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5d9-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a5d9-128">INPUTS</span></span>

## <span data-ttu-id="0a5d9-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a5d9-129">OUTPUTS</span></span>

### <span data-ttu-id="0a5d9-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="0a5d9-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="0a5d9-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a5d9-131">NOTES</span></span>

<span data-ttu-id="0a5d9-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0a5d9-132">ALIASES</span></span>

## <span data-ttu-id="0a5d9-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a5d9-133">RELATED LINKS</span></span>

