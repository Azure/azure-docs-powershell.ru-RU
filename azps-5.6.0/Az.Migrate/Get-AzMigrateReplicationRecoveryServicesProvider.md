---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: 2e890de56cdcf0ac2b17853b10629a58fce6c3b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982835"
---
# <span data-ttu-id="9052d-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="9052d-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="9052d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9052d-102">SYNOPSIS</span></span>
<span data-ttu-id="9052d-103">Сведения о зарегистрированных поставщиках услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="9052d-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="9052d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9052d-104">SYNTAX</span></span>

### <span data-ttu-id="9052d-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9052d-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9052d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="9052d-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9052d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9052d-107">DESCRIPTION</span></span>
<span data-ttu-id="9052d-108">Сведения о зарегистрированных поставщиках услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="9052d-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="9052d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9052d-109">EXAMPLES</span></span>

### <span data-ttu-id="9052d-110">Пример 1. Все поставщики в сейфе</span><span class="sxs-lookup"><span data-stu-id="9052d-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="9052d-111">Перечислить все.</span><span class="sxs-lookup"><span data-stu-id="9052d-111">List all.</span></span>

## <span data-ttu-id="9052d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9052d-112">PARAMETERS</span></span>

### <span data-ttu-id="9052d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9052d-113">-DefaultProfile</span></span>
<span data-ttu-id="9052d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9052d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9052d-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="9052d-115">-FabricName</span></span>
<span data-ttu-id="9052d-116">Имя ткань.</span><span class="sxs-lookup"><span data-stu-id="9052d-116">Fabric name.</span></span>

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

### <span data-ttu-id="9052d-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="9052d-117">-ProviderName</span></span>
<span data-ttu-id="9052d-118">Имя поставщика услуг восстановления</span><span class="sxs-lookup"><span data-stu-id="9052d-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="9052d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9052d-119">-ResourceGroupName</span></span>
<span data-ttu-id="9052d-120">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="9052d-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="9052d-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9052d-121">-ResourceName</span></span>
<span data-ttu-id="9052d-122">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="9052d-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="9052d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9052d-123">-SubscriptionId</span></span>
<span data-ttu-id="9052d-124">Azure Subscription Id, в котором был создан проект переноса.</span><span class="sxs-lookup"><span data-stu-id="9052d-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="9052d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9052d-125">CommonParameters</span></span>
<span data-ttu-id="9052d-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9052d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9052d-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9052d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9052d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9052d-128">INPUTS</span></span>

## <span data-ttu-id="9052d-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9052d-129">OUTPUTS</span></span>

### <span data-ttu-id="9052d-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="9052d-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="9052d-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9052d-131">NOTES</span></span>

<span data-ttu-id="9052d-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9052d-132">ALIASES</span></span>

## <span data-ttu-id="9052d-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9052d-133">RELATED LINKS</span></span>

