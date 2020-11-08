---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250068"
---
# <span data-ttu-id="6a96c-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="6a96c-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="6a96c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6a96c-102">SYNOPSIS</span></span>
<span data-ttu-id="6a96c-103">Получает подробные сведения о политике репликации.</span><span class="sxs-lookup"><span data-stu-id="6a96c-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="6a96c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6a96c-104">SYNTAX</span></span>

### <span data-ttu-id="6a96c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6a96c-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6a96c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="6a96c-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6a96c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a96c-107">DESCRIPTION</span></span>
<span data-ttu-id="6a96c-108">Получает подробные сведения о политике репликации.</span><span class="sxs-lookup"><span data-stu-id="6a96c-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="6a96c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6a96c-109">EXAMPLES</span></span>

### <span data-ttu-id="6a96c-110">Пример 1: получение всех политик в хранилище</span><span class="sxs-lookup"><span data-stu-id="6a96c-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="6a96c-111">Получить все политики.</span><span class="sxs-lookup"><span data-stu-id="6a96c-111">Get all policies.</span></span>

### <span data-ttu-id="6a96c-112">Пример 2: получение определенной политики</span><span class="sxs-lookup"><span data-stu-id="6a96c-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="6a96c-113">Получить конкретное значение.</span><span class="sxs-lookup"><span data-stu-id="6a96c-113">Get a specific one.</span></span>

## <span data-ttu-id="6a96c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6a96c-114">PARAMETERS</span></span>

### <span data-ttu-id="6a96c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a96c-115">-DefaultProfile</span></span>
<span data-ttu-id="6a96c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a96c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a96c-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="6a96c-117">-PolicyName</span></span>
<span data-ttu-id="6a96c-118">Имя политики репликации.</span><span class="sxs-lookup"><span data-stu-id="6a96c-118">Replication policy name.</span></span>

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

### <span data-ttu-id="6a96c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a96c-119">-ResourceGroupName</span></span>
<span data-ttu-id="6a96c-120">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="6a96c-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="6a96c-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6a96c-121">-ResourceName</span></span>
<span data-ttu-id="6a96c-122">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="6a96c-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="6a96c-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6a96c-123">-SubscriptionId</span></span>
<span data-ttu-id="6a96c-124">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="6a96c-124">The subscription Id.</span></span>

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

### <span data-ttu-id="6a96c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a96c-125">CommonParameters</span></span>
<span data-ttu-id="6a96c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6a96c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a96c-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a96c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a96c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6a96c-128">INPUTS</span></span>

## <span data-ttu-id="6a96c-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a96c-129">OUTPUTS</span></span>

### <span data-ttu-id="6a96c-130">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="6a96c-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="6a96c-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6a96c-131">NOTES</span></span>

<span data-ttu-id="6a96c-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="6a96c-132">ALIASES</span></span>

## <span data-ttu-id="6a96c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a96c-133">RELATED LINKS</span></span>

