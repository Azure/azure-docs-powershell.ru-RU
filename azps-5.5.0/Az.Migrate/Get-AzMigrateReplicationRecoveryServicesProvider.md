---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: e706e9eb21f601ed1a266faa0afb888297f17fdb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224225"
---
# <span data-ttu-id="1cfde-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1cfde-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="1cfde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cfde-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfde-103">Сведения о зарегистрированных поставщиках услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="1cfde-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="1cfde-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1cfde-104">SYNTAX</span></span>

### <span data-ttu-id="1cfde-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1cfde-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1cfde-106">Получить</span><span class="sxs-lookup"><span data-stu-id="1cfde-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cfde-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cfde-107">DESCRIPTION</span></span>
<span data-ttu-id="1cfde-108">Подробные сведения о зарегистрированных поставщиках услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="1cfde-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="1cfde-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1cfde-109">EXAMPLES</span></span>

### <span data-ttu-id="1cfde-110">Пример 1. Все поставщики в сейфе</span><span class="sxs-lookup"><span data-stu-id="1cfde-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="1cfde-111">Перечислить все.</span><span class="sxs-lookup"><span data-stu-id="1cfde-111">List all.</span></span>

## <span data-ttu-id="1cfde-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cfde-112">PARAMETERS</span></span>

### <span data-ttu-id="1cfde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfde-113">-DefaultProfile</span></span>
<span data-ttu-id="1cfde-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cfde-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cfde-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="1cfde-115">-FabricName</span></span>
<span data-ttu-id="1cfde-116">Имя ткань.</span><span class="sxs-lookup"><span data-stu-id="1cfde-116">Fabric name.</span></span>

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

### <span data-ttu-id="1cfde-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="1cfde-117">-ProviderName</span></span>
<span data-ttu-id="1cfde-118">Имя поставщика услуг восстановления</span><span class="sxs-lookup"><span data-stu-id="1cfde-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="1cfde-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cfde-119">-ResourceGroupName</span></span>
<span data-ttu-id="1cfde-120">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="1cfde-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="1cfde-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1cfde-121">-ResourceName</span></span>
<span data-ttu-id="1cfde-122">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="1cfde-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="1cfde-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1cfde-123">-SubscriptionId</span></span>
<span data-ttu-id="1cfde-124">Azure Subscription Id, в котором был создан проект переноса.</span><span class="sxs-lookup"><span data-stu-id="1cfde-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="1cfde-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfde-125">CommonParameters</span></span>
<span data-ttu-id="1cfde-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cfde-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfde-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cfde-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfde-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cfde-128">INPUTS</span></span>

## <span data-ttu-id="1cfde-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1cfde-129">OUTPUTS</span></span>

### <span data-ttu-id="1cfde-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1cfde-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="1cfde-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1cfde-131">NOTES</span></span>

<span data-ttu-id="1cfde-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1cfde-132">ALIASES</span></span>

## <span data-ttu-id="1cfde-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cfde-133">RELATED LINKS</span></span>

