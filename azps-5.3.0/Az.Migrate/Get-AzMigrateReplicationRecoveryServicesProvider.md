---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505087"
---
# <span data-ttu-id="cca3a-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="cca3a-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="cca3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca3a-102">SYNOPSIS</span></span>
<span data-ttu-id="cca3a-103">Подробные сведения о зарегистрированных поставщиках услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="cca3a-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="cca3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cca3a-104">SYNTAX</span></span>

### <span data-ttu-id="cca3a-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cca3a-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cca3a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="cca3a-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cca3a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cca3a-107">DESCRIPTION</span></span>
<span data-ttu-id="cca3a-108">Подробные сведения о зарегистрированных поставщиках услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="cca3a-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="cca3a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cca3a-109">EXAMPLES</span></span>

### <span data-ttu-id="cca3a-110">Пример 1. Все поставщики в сейфе</span><span class="sxs-lookup"><span data-stu-id="cca3a-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="cca3a-111">Перечислить все.</span><span class="sxs-lookup"><span data-stu-id="cca3a-111">List all.</span></span>

## <span data-ttu-id="cca3a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cca3a-112">PARAMETERS</span></span>

### <span data-ttu-id="cca3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca3a-113">-DefaultProfile</span></span>
<span data-ttu-id="cca3a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cca3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cca3a-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="cca3a-115">-FabricName</span></span>
<span data-ttu-id="cca3a-116">Имя ткань.</span><span class="sxs-lookup"><span data-stu-id="cca3a-116">Fabric name.</span></span>

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

### <span data-ttu-id="cca3a-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="cca3a-117">-ProviderName</span></span>
<span data-ttu-id="cca3a-118">Имя поставщика услуг восстановления</span><span class="sxs-lookup"><span data-stu-id="cca3a-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="cca3a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca3a-119">-ResourceGroupName</span></span>
<span data-ttu-id="cca3a-120">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cca3a-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="cca3a-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cca3a-121">-ResourceName</span></span>
<span data-ttu-id="cca3a-122">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cca3a-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="cca3a-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cca3a-123">-SubscriptionId</span></span>
<span data-ttu-id="cca3a-124">ИД подписки.</span><span class="sxs-lookup"><span data-stu-id="cca3a-124">The subscription Id.</span></span>

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

### <span data-ttu-id="cca3a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca3a-125">CommonParameters</span></span>
<span data-ttu-id="cca3a-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cca3a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca3a-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cca3a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca3a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cca3a-128">INPUTS</span></span>

## <span data-ttu-id="cca3a-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cca3a-129">OUTPUTS</span></span>

### <span data-ttu-id="cca3a-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="cca3a-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="cca3a-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cca3a-131">NOTES</span></span>

<span data-ttu-id="cca3a-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cca3a-132">ALIASES</span></span>

## <span data-ttu-id="cca3a-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cca3a-133">RELATED LINKS</span></span>

