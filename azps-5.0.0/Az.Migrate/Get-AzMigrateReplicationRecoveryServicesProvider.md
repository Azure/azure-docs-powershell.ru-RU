---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250061"
---
# <span data-ttu-id="8e574-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8e574-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="8e574-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e574-102">SYNOPSIS</span></span>
<span data-ttu-id="8e574-103">Получает подробные сведения о зарегистрированном поставщике служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="8e574-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="8e574-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e574-104">SYNTAX</span></span>

### <span data-ttu-id="8e574-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e574-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e574-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8e574-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e574-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e574-107">DESCRIPTION</span></span>
<span data-ttu-id="8e574-108">Получает подробные сведения о зарегистрированном поставщике служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="8e574-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="8e574-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e574-109">EXAMPLES</span></span>

### <span data-ttu-id="8e574-110">Пример 1: получение всех поставщиков в хранилище</span><span class="sxs-lookup"><span data-stu-id="8e574-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="8e574-111">Список всех.</span><span class="sxs-lookup"><span data-stu-id="8e574-111">List all.</span></span>

## <span data-ttu-id="8e574-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e574-112">PARAMETERS</span></span>

### <span data-ttu-id="8e574-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e574-113">-DefaultProfile</span></span>
<span data-ttu-id="8e574-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e574-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e574-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="8e574-115">-FabricName</span></span>
<span data-ttu-id="8e574-116">Имя структуры.</span><span class="sxs-lookup"><span data-stu-id="8e574-116">Fabric name.</span></span>

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

### <span data-ttu-id="8e574-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="8e574-117">-ProviderName</span></span>
<span data-ttu-id="8e574-118">Имя поставщика служб восстановления</span><span class="sxs-lookup"><span data-stu-id="8e574-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="8e574-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e574-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e574-120">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="8e574-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="8e574-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8e574-121">-ResourceName</span></span>
<span data-ttu-id="8e574-122">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="8e574-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="8e574-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e574-123">-SubscriptionId</span></span>
<span data-ttu-id="8e574-124">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="8e574-124">The subscription Id.</span></span>

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

### <span data-ttu-id="8e574-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e574-125">CommonParameters</span></span>
<span data-ttu-id="8e574-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e574-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e574-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e574-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e574-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e574-128">INPUTS</span></span>

## <span data-ttu-id="8e574-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e574-129">OUTPUTS</span></span>

### <span data-ttu-id="8e574-130">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="8e574-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="8e574-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e574-131">NOTES</span></span>

<span data-ttu-id="8e574-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="8e574-132">ALIASES</span></span>

## <span data-ttu-id="8e574-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e574-133">RELATED LINKS</span></span>

