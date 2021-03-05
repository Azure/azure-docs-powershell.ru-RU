---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 25106d6facb65346360bf7c78b7cbef27fc9a517
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982936"
---
# <span data-ttu-id="d4a33-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="d4a33-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="d4a33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4a33-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a33-103">Подробные сведения о структуре восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a33-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="d4a33-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4a33-104">SYNTAX</span></span>

### <span data-ttu-id="d4a33-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4a33-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d4a33-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d4a33-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d4a33-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4a33-107">DESCRIPTION</span></span>
<span data-ttu-id="d4a33-108">Подробные сведения о структуре восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a33-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="d4a33-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4a33-109">EXAMPLES</span></span>

### <span data-ttu-id="d4a33-110">Пример 1. Получить все ткань по названию группы ресурсов и хранилища</span><span class="sxs-lookup"><span data-stu-id="d4a33-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="d4a33-111">Получить все ткань в группе и хранилище ресурсов</span><span class="sxs-lookup"><span data-stu-id="d4a33-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="d4a33-112">Пример 2. Получить материал по группе ресурсов, имени сейфа и имени ткань</span><span class="sxs-lookup"><span data-stu-id="d4a33-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="d4a33-113">Получить определенный материал</span><span class="sxs-lookup"><span data-stu-id="d4a33-113">Get a specific fabric</span></span>

## <span data-ttu-id="d4a33-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4a33-114">PARAMETERS</span></span>

### <span data-ttu-id="d4a33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a33-115">-DefaultProfile</span></span>
<span data-ttu-id="d4a33-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a33-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a33-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="d4a33-117">-FabricName</span></span>
<span data-ttu-id="d4a33-118">Имя ткань.</span><span class="sxs-lookup"><span data-stu-id="d4a33-118">Fabric name.</span></span>

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

### <span data-ttu-id="d4a33-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a33-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4a33-120">Имя группы ресурсов, в которой находится хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d4a33-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="d4a33-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d4a33-121">-ResourceName</span></span>
<span data-ttu-id="d4a33-122">Имя хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d4a33-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="d4a33-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4a33-123">-SubscriptionId</span></span>
<span data-ttu-id="d4a33-124">Azure Subscription Id, в котором был создан проект переноса.</span><span class="sxs-lookup"><span data-stu-id="d4a33-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d4a33-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a33-125">CommonParameters</span></span>
<span data-ttu-id="d4a33-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a33-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a33-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4a33-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a33-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4a33-128">INPUTS</span></span>

## <span data-ttu-id="d4a33-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4a33-129">OUTPUTS</span></span>

### <span data-ttu-id="d4a33-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span><span class="sxs-lookup"><span data-stu-id="d4a33-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="d4a33-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4a33-131">NOTES</span></span>

<span data-ttu-id="d4a33-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d4a33-132">ALIASES</span></span>

## <span data-ttu-id="d4a33-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4a33-133">RELATED LINKS</span></span>

